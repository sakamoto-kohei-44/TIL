require 'rails_helper'

Rspec.describe "AdminArticlesPreview", type: :system do
  let(:admin) { create :user,  :admin }
  describe '記事作成画面で画像ブロックを追加'
    context '画像ファイルをアップロードせずにプレビューページを閲覧できる'
      it '正常に表示される'
        login(admin) #「管理者(admin)としてログインする」っていう動作
        click_link '記事'
        visit admin_artcles_path
        click_link '新規作成'
        visit admin_artcles
        ddd
